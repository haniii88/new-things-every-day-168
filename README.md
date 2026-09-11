function dailyLog168() {
  const results = [
    { name: "Coding", score: 92 },
    { name: "Reading", score: 78 },
    { name: "Exercise", score: 85 },
    { name: "Learning", score: 95 }
  ];

  const totalScore = results.reduce(
    (sum, result) => sum + result.score,
    0
  );

  const bestResult = results.reduce((best, result) =>
    result.score > best.score ? result : best
  );

  const report = {
    date: new Date().toISOString().split("T")[0],
    totalScore,
    averageScore: (totalScore / results.length).toFixed(1),
    bestActivity: bestResult.name,
    bestScore: bestResult.score
  };

  console.log("Daily Score Report:", report);
}

dailyLog168();
